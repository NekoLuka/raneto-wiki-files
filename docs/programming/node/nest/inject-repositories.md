### Inject repositories

### Example:

```ts
@Injectable()
export class UsersService {
  constructor(@InjectRepository(User) private userRepo: Repository<User>) {}
}
```
